---
title: Verwalten von Druckern in einem MED-V-Arbeitsbereich
description: Verwalten von Druckern in einem MED-V-Arbeitsbereich
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811563"
---
# Verwalten von Druckern in einem MED-V-Arbeitsbereich


In Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 bietet die Druckerumleitung Endbenutzern eine konsistente Druckfunktionalität zwischen dem virtuellen Med-v-Computer und dem Hostcomputer.

Dieses Thema enthält Informationen zum Verwalten des Druckvorgangs in einem MED-V-Arbeitsbereich.

## Verwalten von Druckern in MED-V-Arbeitsbereichen


In den meisten Fällen verarbeitet MED-V die Druckerumleitung automatisch. Nach Abschluss der erstmaligen Einrichtung identifiziert Med-v alle auf dem Host installierten Netzwerkdrucker, ruft die entsprechenden Treiber vom Netzwerkdruckserver ab und installiert die entsprechenden Treiber im Med-v-Arbeitsbereich, wenn Sie gefunden wurden. Nachdem alle Treiber gefunden und installiert wurden, startet Med-v den Med-v-Arbeitsbereich neu. Erst nachdem der MED-V-Arbeitsbereich neu gestartet wurde, sind die Host Drucker vorhanden und für den Gast verfügbar, in der Regel in wenigen Minuten.

**Hinweis**  Wenn Anwendungen im MED-V-Arbeitsbereich ausgeführt werden, wird der Endbenutzer aufgefordert, den Neustart fortzusetzen oder zu einem späteren Zeitpunkt zu verschieben. Wenn keine Anwendungen ausgeführt werden, ist der Neustart automatisch und wird dem Endbenutzer nicht angezeigt.

 

Jedes Mal, wenn MED-V neu gestartet wird, überprüft es, ob neue Drucker auf dem Host installiert sind, und ruft, falls gefunden, die entsprechenden Treiber vom Netzwerkdruckserver ab und installiert Sie auf dem Gast. Med-v startet den Med-v-Arbeitsbereich so neu, wie wenn die erstmalige Einrichtung abgeschlossen wurde.

**Wichtig**  Nachdem die relevanten Treiber auf dem Gast installiert wurden, werden die Drucker erst nach dem Neustart auf dem Gast sichtbar.

 

Wenn ein Treiber zu einem beliebigen Zeitpunkt nicht gefunden oder installiert werden kann, muss er manuell auf dem Gast installiert sein, damit der Netzwerkdrucker für den Endbenutzer zur Verfügung steht.

Die folgende Liste enthält einige zusätzliche Anleitungen:

In **MED-V werden nur Netzwerkdrucker verwaltet**. Treiber für Drucker, die lokal auf dem Host installiert sind, werden auf dem Gast nicht automatisch installiert.

**In MED-V werden nur Druckertreiber installiert, wenn Sie auf dem Druckserver gefunden**werden. Wenn Sie nicht gefunden werden, müssen die Druckertreiber manuell installiert werden.

**Drucker, die manuell auf dem Gast installiert sind, sind für den Host nicht zugänglich**. Standardmäßig unterstützt MED-V nur die Druckerumleitung vom Gast zum Host.

**Warnung**  Wenn ein Drucker manuell auf dem Gast installiert ist und der Drucker später auf dem Host installiert ist, ist das Ergebnis, dass der Drucker zwei Mal im Gast installiert ist. Um dieses Problem zu vermeiden, empfiehlt es sich, die Druckerumleitung nur auf eine Art und Weise zu verwalten: entweder deaktivieren Sie die Umleitung, und installieren Sie Drucker manuell auf dem Gast, oder aktivieren Sie die Umleitung, und installieren Sie Drucker nicht manuell auf dem Gast.

 

## Verwandte Themen


[Verwalten von MED-V-Arbeitsbereichseinstellungen](manage-med-v-workspace-settings.md)

 

 





