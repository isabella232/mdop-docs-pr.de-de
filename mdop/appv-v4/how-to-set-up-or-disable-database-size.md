---
title: So richten Sie die Datenbankgröße ein oder deaktivieren Sie sie
description: So richten Sie die Datenbankgröße ein oder deaktivieren Sie sie
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806756"
---
# So richten Sie die Datenbankgröße ein oder deaktivieren Sie sie


Mit den folgenden Verfahren können Sie in der Application Virtualization Server-Verwaltungskonsole die Größe (in MB) der Application Virtualization System-Nutzung angeben, die in der Datenbank gespeichert werden soll.

Wenn die Größe der gespeicherten Daten 95% (das höchst Wasserzeichen) des angegebenen Grenzwerts erreicht, löscht das System 10% der Nutzungsdaten, wobei 85% der Daten übrig sind. Paket-und Anwendungs Nutzungsdaten werden gelöscht. Wenn die Datenbank groß genug ist und sich dem hohen Wasserzeichen nähert, wird eine Warnmeldung an das SQL Server-Protokoll gesendet, um Sie darüber zu informieren, dass dieser Grenzwert erreicht wurde. Diese Warnung ist erforderlich, da sich die Bereinigungsaktion auf die Ausgabe der Berichte auswirken kann. Darüber hinaus können Sie entscheiden, ob Sie die maximale Datenbankgröße erhöhen, die Anzahl der Monate für die Aufbewahrung der Nutzungsdaten verringern oder den Protokolliergrad reduzieren müssen.

**Hinweis**  Die Optionen " **keine Größe begrenzen** " und " **alle Verwendung beibehalten** " werden bereitgestellt, damit Sie die Verwendungsberichterstattung und die Datenbankbereinigung deaktivieren können. Durch Auswahl dieser Elemente wird auch das Datenbanktransaktionsprotokoll bereinigt. (Alle übernommenen Microsoft SQL Server-Transaktionen werden aus dem Datenbankprotokoll entfernt.)

 

**So richten Sie die Datenbankgröße ein**

1.  Klicken Sie im linken Bereich mit der rechten Maustaste auf den Knoten Application Virtualization System, und wählen Sie **Systemoptionen**aus.

2.  Wählen Sie die Registerkarte **Datenbank** aus.

3.  Aktivieren Sie das Optionsfeld **maximale Datenbankgröße (MB)** oder **keine Größenbeschränkung** .

4.  Wenn Sie sich entscheiden, eine Datenbankgröße anzugeben, empfehlen bewährte Methoden, eine Zahl zwischen 512 und 4096 MB einzugeben. Die Standardgröße ist 1024 MB, und wenn Sie die Datenbankgröße erhöhen müssen, ist der Maximalwert, den Sie eingeben können, 2.147.483.647. Wenn Sie **keine Größenbeschränkung**auswählen, wird die Datenbank so lange vergrößert, bis Sie den Grenzwert für die Datenträgergröße erreicht hat.

5.  Klicken Sie auf über **nehmen** oder **OK**.

**So deaktivieren Sie die Größenbeschränkungen für Datenbanken**

1.  Klicken Sie im **Bereich** Bereich mit der rechten Maustaste auf den Knoten Application Virtualization System, und wählen Sie **Systemoptionen**aus.

2.  Wählen Sie die Registerkarte **Datenbank** aus.

3.  Wählen Sie die Optionsfelder **keine Größenbeschränkung** und **alle Verwendung beibehalten** aus.

4.  Klicken Sie auf über **nehmen** oder **OK**.

## Verwandte Themen


[So passen Sie ein Application Virtualization System in der Server Management Console an](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[So richten Sie die Verwendungsberichterstellung ein oder deaktivieren Sie sie](how-to-set-up-or-disable-usage-reporting.md)

 

 





