---
title: Verbessern der Sicherheit während der App-V-Sequenzierung
description: Verbessern der Sicherheit während der App-V-Sequenzierung
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806675"
---
# Verbessern der Sicherheit während der App-V-Sequenzierung


Verpackungsanwendungen für die Sequenzierung sind die größte fortlaufende Aufgabe in einer App-V-Infrastruktur. Da es sich um eine laufende Aufgabe handelt, sollten Sie sorgfältig die Erstellung von Richtlinien und Verfahren für die Sequenzierung von Anwendungen in Frage stellen. In App-v 4.5 können Sie während der Sequenzierung Zugriffssteuerungslisten (ACLs) für die Dateiressourcen der virtualisierten Anwendung aufzeichnen.

## Virenscan auf dem Sequenzer


Es wird empfohlen, die Scansoftware auf dem Sequenzcomputer zu installieren und den Computer dann auf Viren und Malware zu überprüfen. Deaktivieren Sie die Scansoftware, einschließlich aller Antivirus-und Malware Erkennungssoftware, auf dem Sequenzcomputer, bevor Sie alle Anwendungen sequenzieren, nachdem der Sequenzcomputer gescannt und virenfrei oder Malware freigegeben wurde. Dies beschleunigt den Sequenzierungsprozess und verhindert, dass die Scansoftware Komponenten während der Sequenzierung erkannt und im virtuellen Anwendungspaket enthalten sind.

## Aufzeichnen von ACLs für Dateien (NTFS)


Der Sequencer zeichnet NTFS-Berechtigungen (ACLs) für die Dateien auf, die während der Installationsphase der Sequenz Überwachung überwacht werden. (Vor der Veröffentlichung von App-v 4.5 wurden ACLs nicht als Teil des Sequenz Prozesses erfasst.) Mit diesem neuen Feature können bestimmte Anwendungen für Benutzer mit einer geringen Berechtigungsstufe ausgeführt werden, für die normalerweise Administratorrechte erforderlich sind.

Dieses Feature ermöglicht es dem Sequenz Ingenieur auch, die vom Hersteller identifizierten Sicherheitseinstellungen zu erfassen. Wenn die vom Hersteller empfohlenen Einstellungen nicht angewendet werden, kann die Anwendung für Angriffe oder Missbrauch durch die Benutzer geöffnet bleiben. Informationen dazu, ob Sie eine Anwendung mit geöffneten ACLs bereitstellen sollten, finden Sie unter Anwendungssupport Gruppe oder Softwarehersteller.

**Wichtig**  Obwohl der Sequencer die NTFS-ACLs erfasst, während die Installationsphase der Sequenzierung überwacht wird, werden die ACLs für die Registrierung nicht erfasst. Benutzer haben vollständigen Zugriff auf alle Registrierungsschlüssel für virtuelle Anwendungen mit Ausnahme der Dienste. Wenn ein Benutzer jedoch die Registrierung einer virtuellen Anwendung ändert, wird diese Änderung an einem bestimmten Speicherort ( `uservol_sftfs_v1.pkg` ) gespeichert und wirkt sich nicht auf andere Benutzer aus.

 

Während der Installationsphase kann ein Sequenz Ingenieur die Standardberechtigungen der Dateien bei Bedarf ändern. Nach Abschluss des Sequenz Prozesses, aber vor dem Speichern des Pakets, kann der Sequenz Ingenieur dann Sicherheitsdeskriptoren erzwingen, die während der Installationsphase aufgezeichnet wurden. Es ist eine bewährte Methode, Sicherheitsbeschreibungen zu erzwingen, wenn keine andere Lösung die ordnungsgemäße Ausführung der Anwendung ermöglicht.

 

 





