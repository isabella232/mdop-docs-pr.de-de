---
title: Versionshinweise für Microsoft Advanced Group Policy Management 4.0
description: Versionshinweise für Microsoft Advanced Group Policy Management 4.0
author: dansimp
ms.assetid: 44c19e61-c8e8-48aa-a2c2-20396d14d5bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c4a279893d4da4121e422af99e7c1708a0126b4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808288"
---
# Versionshinweise für Microsoft Advanced Group Policy Management 4.0


Oktober2009

## Informationen zur erweiterten Microsoft-Gruppenrichtlinienverwaltung 4,0


Microsoft Advanced Group Policy Management (AGPM) 4,0 erweitert die Funktionen der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC). AGPM bietet umfassende Änderungssteuerung und verbesserte Verwaltung von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs).

Die folgenden Dokumente können Ihnen bei den ersten Schritten mit AGPM 4,0 helfen.

-   Eine Übersicht über die Funktionen von AGPM finden Sie unter [Übersicht über die Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkID=162671) ( https://go.microsoft.com/fwlink/?LinkID=162671) .

-   Informationen dazu, wie AGPM 4,0 von AGPM 3,0 abweicht, finden Sie unter [Neuerungen in AGPM 4,0](https://go.microsoft.com/fwlink/?LinkId=160058) ( https://go.microsoft.com/fwlink/?LinkId=160058) .

-   Informationen dazu, wie Sie feststellen können, ob AGPM 4,0, AGPM 3,0 oder AGPM 2,5 für Ihre Umgebung geeignet ist, finden Sie unter [Auswählen der zu installierenden AGPM-Version](https://go.microsoft.com/fwlink/?LinkId=145981) ( https://go.microsoft.com/fwlink/?LinkId=145981) .

-   Grundlegende Anleitungen zum Installieren von AGPM und eines Beispielszenarios für die Verwendung von AGPM finden Sie unter [schrittweise Anleitung für Microsoft Advanced Group Policy Management 4,0](https://go.microsoft.com/fwlink/?LinkID=153505) ( https://go.microsoft.com/fwlink/?LinkID=153505) . Dieser Leitfaden dient in erster Linie dazu, Evaluatoren und Erstbenutzern zu helfen.

-   Informationen zum Upgrade von einer früheren Version von AGPM oder ausführliche Anleitungen zum Planen der Bereitstellung von AGPM in Ihrer Organisation finden Sie im [Planungshandbuch für Microsoft Advanced Group Policy Management 4,0](https://go.microsoft.com/fwlink/?LinkID=156883) ( https://go.microsoft.com/fwlink/?LinkID=156883) .

-   Informationen zum Verwenden von AGPM zum Ausführen bestimmter Aufgaben finden Sie in der Hilfe zur erweiterten Gruppenrichtlinienverwaltung 4,0, die auch auf TechNet als [Betriebshandbuch für AGPM 4,0](https://go.microsoft.com/fwlink/?LinkId=159872) ( https://go.microsoft.com/fwlink/?LinkId=159872) .

## Weitere Informationen


Weitere Informationen zu AGPM finden Sie unter den folgenden Themen:

-   [Erweiterte TechNet-Bibliothek für Gruppenrichtlinienverwaltung](https://go.microsoft.com/fwlink/?LinkID=146846) (https://go.microsoft.com/fwlink/?LinkID=146846)

-   [Microsoft Desktop Optimization Pack-TechCenter](https://go.microsoft.com/fwlink/?LinkId=159870) (https://www.microsoft.com/technet/mdop)

-   [Gruppenrichtlinien-TechCenter](https://go.microsoft.com/fwlink/?LinkId=145531) (https://www.microsoft.com/gp)

## Abgeben von Feedback


Sie können Feedback oder Fragen zu AGPM im [Gruppenrichtlinien Forum](https://go.microsoft.com/fwlink/?LinkId=145532) Posten ( https://go.microsoft.com/fwlink/?LinkId=145532) .

## Bekannte Probleme mit AGPM 4,0


### Befehl ' aus Produktion importieren ' importiert keine Einstellungen in ein GPO, das ausgecheckt ist.

Wenn Sie ein GPO in der Produktionsumgebung bearbeiten, müssen Sie das Gruppenrichtlinienobjekt aus der Produktion importieren, um das Gruppenrichtlinienobjekt im Offline Archiv zu aktualisieren. Mit dem Befehl " **aus Produktion importieren** " können Sie eine endgültige Produktionssicherung durchführen, bevor Sie die Bearbeitung abgeschlossen haben, sodass Sie bei Bedarf ein Rollback zur Produktionssicherung durchführen können.

Wenn das Gruppenrichtlinienobjekt ausgecheckt ist, wenn Sie den Befehl **aus Produktion importieren** ausführen, werden die Produktionsänderungen nicht in die ausgecheckte Version des Gruppenrichtlinienobjekts übernommen. Die importierte Version des Gruppenrichtlinienobjekts wird jedoch dem Verlauf des Gruppenrichtlinienobjekts hinzugefügt, obwohl diese Version nicht zur Bearbeitung zur Verfügung steht. Wenn das Gruppenrichtlinienobjekt eingecheckt ist, ersetzt diese Version die importierte Version im Archiv, aber beide sind im Verlauf des Gruppenrichtlinienobjekts verfügbar.

**Problemumgehung:** Stellen Sie sicher, dass das Gruppenrichtlinienobjekt eingecheckt ist, bevor Sie es aus Production importieren. Wenn das Gruppenrichtlinienobjekt nicht eingecheckt wurde, bevor Sie es importiert haben, können Sie den Befehl **Auschecken rückgängig** verwenden, um Ihre Änderungen zu verwerfen und die Version des Gruppenrichtlinienobjekts zurückzusetzen, das Sie aus der Produktionsumgebung importiert haben.

### Ausgecheckte GPOs können in einer Umgebung mit einer Active Directory-Topologie mit mehreren Standorten nicht für mehrere Minuten bearbeitet werden

AGPM verwendet ein Client/Server-Modell. Der AGPM-Server und der AGPM-Client bestimmen jeweils seinen eigenen nächstgelegenen Domänencontroller für Gruppenrichtlinienvorgänge. Wenn Sie ein GPO mithilfe eines AGPM-Clients Auschecken, überprüft der AGPM-Server das Gruppenrichtlinienobjekt aus dem Offline Archiv in einen temporären Ordner im Ordner "SYSVOL".

Wenn sich der AGPM-Server und der AGPM-Client an verschiedenen Standorten befinden, ist das temporäre ausgecheckte Gruppenrichtlinienobjekt auf dem Domänencontroller der lokalen Website für mehrere Minuten oder bis zu 30 Minuten aufgrund der SYSVOL-Replikationswartezeit möglicherweise nicht vorhanden. In diesem Fall können Sie das ausgecheckte Gruppenrichtlinienobjekt nicht mit der GPMC auf einem AGPM-Client bearbeiten, bis die SYSVOL-Replikation des ausgecheckten Gruppenrichtlinienobjekts stattgefunden hat.

**Problemumgehung:** Als bewährte Methode sollten Sie AGPM-Clients am gleichen Standort wie der AGPM-Server positionieren, mit dem Sie eine Verbindung herstellen, damit Sie nicht warten müssen, bis die SYSVOL-Replikation erfolgt, bevor Sie ein ausgechecktes Gruppenrichtlinienobjekt bearbeiten können.

### AGPM kann den Sicherungs Grenzwert nicht lesen, wenn Ihr Konto nicht über die Berechtigungen für das Archiv verfügt

Wenn Sie sich bei einem AGPM-Client mit einem Konto anmelden, dem keine Berechtigungen für das AGPM-Archiv zugewiesen wurden, starten Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC), und klicken Sie dann auf **Steuerelement ändern**, wenn Sie die folgende Fehlermeldung erhalten.

``` syntax
Failed to read backup purge limit for this domain. 

The following error occurred: 
You do not have sufficient permissions to perform this operation. 
Microsoft.Agpm.AccessDeniedException (80070005)
```

**Problemumgehung:** Wenden Sie sich an einen AGPM-Administrator (Vollzugriff), und fordern Sie die Stellvertretung des Zugriffs auf AGPM für Ihr Konto an. Wenn Sie ein AGPM-Administrator sind, melden Sie sich mit einem Konto an, dem die AGPM-Administratorrolle zugewiesen ist, damit Sie den Zugriff für das zusätzliche Konto delegieren können. Weitere Informationen finden Sie in der Hilfe zu AGPM unter "Delegieren des Zugriffs auf das Archiv auf Domänenebene".

## Anmerkungen zu dieser Version Copyright-Informationen


Informationen in diesem Dokument, einschließlich URLs und anderen Internet-Website verweisen, können ohne Vorankündigung geändert werden und dienen nur zu Informationszwecken. Das gesamte Risiko der Nutzung oder der Ergebnisse der Verwendung dieses Dokuments verbleibt beim Nutzer, und Microsoft Corporation übernimmt keine Garantien, weder ausdrücklich noch impliziert. Die hier gezeigten Beispiele für Unternehmen, Organisationen, Produkte, Personen und Ereignisse sind fiktiv. Keine Assoziation mit einem wirklichen Unternehmen, einer Organisation, einem Produkt, einer Person oder einem Ereignis ist beabsichtigt oder sollte abgeleitet werden. Die Einhaltung aller anwendbaren Urheberrechtsgesetze obliegt dem Nutzer. Ohne die Rechte unter dem Urheberrecht zu begrenzen, darf kein Teil dieses Dokuments reproduziert, gespeichert oder in ein Retrievalsystem aufgenommen oder in irgendeiner Form oder auf andere Weise (elektronisch, mechanisch, Fotokopieren, aufzeichnen oder auf andere Weise) oder zu einem beliebigen Zweck ohne die ausdrückliche schriftliche Genehmigung der Microsoft Corporation übertragen werden.

Microsoft hat möglicherweise Patente, Patentanmeldungen, Marken, Urheberrechte oder andere Rechte an geistigem Eigentum, die Inhalte dieses Dokuments abdecken. Sofern nicht ausdrücklich in einem schriftlichen Lizenzvertrag von Microsoft vorgesehen, gibt Ihnen die Einrichtung dieses Dokuments keine Lizenz für diese Patente, Marken, Urheberrechte oder sonstiges geistiges Eigentum.



Microsoft, MS-DOS, Windows, Windows Server und Windows Vista sind entweder eingetragene Marken oder Marken von MicrosoftCorporation in den USA und/oder anderen Ländern.

Die Namen der Unternehmen und Produkte, die hierin erwähnt werden, können Marken der jeweiligen Besitzer sein.

 

 





