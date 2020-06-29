---
title: Unterbrochener Betriebsmodus
description: Unterbrochener Betriebsmodus
author: dansimp
ms.assetid: 3f9849ea-ba53-4c68-85d3-87a4218f59c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e9534b93f23b17e5258ef5e2d548eb93213f2f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808866"
---
# Unterbrochener Betriebsmodus


Die Einstellungen für den getrennten Betriebsmodus – Barrierefrei, indem Sie mit der rechten Maustaste auf den Knoten **Application Virtualization** klicken, **Eigenschaften**auswählen und auf die Registerkarte **Konnektivität** klicken – ermöglicht es dem Application Virtualization Desktop Client oder-Client für Remote Desktop Dienste (ehemals Terminal Dienste), Anwendungen auszuführen, die im Dateisystemcache des Clients gespeichert sind, wenn der Client keine Verbindung mit dem Application Virtualization Management Server herstellen kann

Gründe für die fehlerhafte Verbindung mit dem Server sind Serverfehler, Netzwerkausfälle oder die Trennung vom Netzwerk. Wenn ein Fehler auftritt, wechselt der Client automatisch in den getrennten Betrieb. Wenn der Client nach dem Trennen der Verbindung zusätzliche Daten vom Server benötigt, um weiterhin eine Anwendung auszuführen, oder wenn das Timeout des getrennten Vorgangs abgelaufen ist, versucht der Client erneut, eine Verbindung mit dem Server herzustellen. Wenn dieser Verbindungsversuch fehlschlägt, wird die Anwendung beendet.

Standardmäßig ist der getrennte Vorgang aktiviert, und das Timeout ist auf 90 Tage festzulegen. Der Timeoutwert wird als die Anzahl der Tage angegeben, die Sie den unterbrochenen Betriebsmodus begrenzen möchten, und Sie können einen Wert von 1 bis 999 eingeben.

## Verwandte Themen


[So deaktivieren oder ändern Sie Einstellungen für den unterbrochenen Betriebsmodus](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





